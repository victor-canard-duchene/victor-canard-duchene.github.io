import React, { useState, useMemo } from 'react';
import { 
  Check, 
  Plus, 
  Trash2, 
  TrendingUp, 
  Calendar, 
  Zap, 
  Activity, 
  Droplets, 
  BookOpen, 
  Moon, 
  Sun,
  Dumbbell,
  Briefcase,
  Music,
  Heart,
  Coffee,
  RotateCcw
} from 'lucide-react';

// --- Icons & Categories ---
const ICONS = {
  general: Activity,
  health: Heart,
  fitness: Dumbbell,
  water: Droplets,
  learning: BookOpen,
  work: Briefcase,
  mindfulness: Moon,
  creativity: Music,
  morning: Coffee,
};

const COLORS = {
  general: 'bg-slate-500',
  health: 'bg-rose-500',
  fitness: 'bg-orange-500',
  water: 'bg-blue-500',
  learning: 'bg-indigo-500',
  work: 'bg-slate-700',
  mindfulness: 'bg-violet-500',
  creativity: 'bg-pink-500',
  morning: 'bg-amber-500',
};

export default function App() {
  // --- State ---
  // In-memory state for the session
  const [habits, setHabits] = useState([
    { id: 1, title: 'Morning Jog', category: 'fitness', streak: 12, completed: false },
    { id: 2, title: 'Drink 2L Water', category: 'water', streak: 5, completed: true },
    { id: 3, title: 'Read 30 mins', category: 'learning', streak: 3, completed: false },
    { id: 4, title: 'Meditation', category: 'mindfulness', streak: 21, completed: true },
  ]);

  const [isAddModalOpen, setIsAddModalOpen] = useState(false);
  const [newHabitTitle, setNewHabitTitle] = useState('');
  const [newHabitCategory, setNewHabitCategory] = useState('general');

  // --- Derived State (Stats) ---
  const stats = useMemo(() => {
    const total = habits.length;
    const completed = habits.filter(h => h.completed).length;
    const progress = total === 0 ? 0 : Math.round((completed / total) * 100);
    const totalStreak = habits.reduce((acc, curr) => acc + curr.streak, 0);
    
    return { total, completed, progress, totalStreak };
  }, [habits]);

  // --- Actions ---
  const toggleHabit = (id) => {
    setHabits(habits.map(habit => {
      if (habit.id === id) {
        // Simple logic: if checking, increment streak. If unchecking, decrement.
        // In a real app with dates, this would be more complex.
        const newCompleted = !habit.completed;
        return {
          ...habit,
          completed: newCompleted,
          streak: newCompleted ? habit.streak + 1 : Math.max(0, habit.streak - 1)
        };
      }
      return habit;
    }));
  };

  const deleteHabit = (id) => {
    setHabits(habits.filter(h => h.id !== id));
  };

  const resetApp = () => {
    if (window.confirm("Are you sure you want to reset everything? This will remove all habits and start from 0.")) {
      setHabits([]);
    }
  };

  const addHabit = (e) => {
    e.preventDefault();
    if (!newHabitTitle.trim()) return;

    const newHabit = {
      id: Date.now(),
      title: newHabitTitle,
      category: newHabitCategory,
      streak: 0,
      completed: false
    };

    setHabits([...habits, newHabit]);
    setNewHabitTitle('');
    setIsAddModalOpen(false);
  };

  // --- Components ---

  const HabitCard = ({ habit }) => {
    const Icon = ICONS[habit.category] || ICONS.general;
    const colorClass = COLORS[habit.category] || COLORS.general;

    return (
      <div className={`group relative flex items-center justify-between p-4 mb-4 bg-white rounded-2xl border border-slate-100 shadow-sm hover:shadow-md transition-all duration-300 ${habit.completed ? 'opacity-80' : ''}`}>
        
        {/* Left Side: Icon & Info */}
        <div className="flex items-center gap-4 flex-1">
          <div className={`p-3 rounded-xl text-white ${colorClass} shadow-sm transition-transform duration-300 group-hover:scale-105`}>
            <Icon size={20} strokeWidth={2.5} />
          </div>
          <div className="flex flex-col">
            <h3 className={`font-bold text-slate-800 text-lg transition-all ${habit.completed ? 'line-through text-slate-400' : ''}`}>
              {habit.title}
            </h3>
            <div className="flex items-center gap-2 text-xs font-medium text-slate-500 uppercase tracking-wider">
              <span className="flex items-center gap-1">
                <Zap size={12} className="text-amber-500" />
                {habit.streak} Day Streak
              </span>
              <span>•</span>
              <span className="opacity-70">{habit.category}</span>
            </div>
          </div>
        </div>

        {/* Right Side: Actions */}
        <div className="flex items-center gap-3">
          <button 
            onClick={() => deleteHabit(habit.id)}
            className="p-2 text-slate-300 hover:text-rose-500 hover:bg-rose-50 rounded-full transition-colors opacity-0 group-hover:opacity-100 focus:opacity-100"
            aria-label="Delete habit"
          >
            <Trash2 size={18} />
          </button>
          
          <button
            onClick={() => toggleHabit(habit.id)}
            className={`
              relative flex items-center justify-center w-12 h-12 rounded-full transition-all duration-300 ease-out border-2
              ${habit.completed 
                ? 'bg-emerald-500 border-emerald-500 text-white scale-110 shadow-emerald-200 shadow-lg' 
                : 'bg-slate-50 border-slate-200 text-slate-300 hover:border-emerald-400 hover:text-emerald-400'
              }
            `}
          >
            <Check size={24} strokeWidth={3} className={`transition-transform duration-300 ${habit.completed ? 'scale-100' : 'scale-75'}`} />
          </button>
        </div>
      </div>
    );
  };

  const StatCard = ({ icon: Icon, label, value, color }) => (
    <div className="bg-white p-4 rounded-2xl border border-slate-100 shadow-sm flex items-center gap-4 flex-1 min-w-[140px]">
      <div className={`p-3 rounded-xl ${color} bg-opacity-10 text-${color.split('-')[1]}-600`}>
        <Icon size={20} />
      </div>
      <div>
        <p className="text-slate-400 text-xs font-bold uppercase tracking-wider">{label}</p>
        <p className="text-slate-800 text-xl font-black">{value}</p>
      </div>
    </div>
  );

  return (
    <div className="min-h-screen bg-slate-50 font-sans text-slate-900 pb-24 md:pb-10 selection:bg-indigo-100">
      
      {/* --- Header Section --- */}
      <header className="sticky top-0 z-10 bg-white/80 backdrop-blur-md border-b border-slate-200/60">
        <div className="max-w-2xl mx-auto px-6 py-4 flex items-center justify-between">
          <div>
            <h1 className="text-2xl font-black bg-gradient-to-r from-indigo-600 to-violet-600 bg-clip-text text-transparent">
              HabitFlow
            </h1>
            <p className="text-slate-500 text-sm font-medium">
              {new Date().toLocaleDateString('en-US', { weekday: 'long', month: 'long', day: 'numeric' })}
            </p>
          </div>
          <div className="flex items-center gap-3">
            <button 
              onClick={resetApp}
              className="h-10 w-10 rounded-full bg-slate-100 text-slate-500 hover:bg-rose-100 hover:text-rose-500 flex items-center justify-center transition-colors"
              title="Reset All Data"
            >
              <RotateCcw size={18} />
            </button>
            <div className="h-10 w-10 rounded-full bg-indigo-100 text-indigo-600 flex items-center justify-center font-bold text-sm">
              ME
            </div>
          </div>
        </div>
      </header>

      <main className="max-w-2xl mx-auto px-6 py-8">
        
        {/* --- Stats Row --- */}
        <div className="flex flex-wrap gap-4 mb-8">
          <StatCard 
            icon={TrendingUp} 
            label="Completion" 
            value={`${stats.progress}%`} 
            color="bg-emerald-500" 
          />
          <StatCard 
            icon={Zap} 
            label="Total Streak" 
            value={stats.totalStreak} 
            color="bg-amber-500" 
          />
          <StatCard 
            icon={Calendar} 
            label="Active Habits" 
            value={stats.total} 
            color="bg-blue-500" 
          />
        </div>

        {/* --- Progress Bar --- */}
        <div className="mb-10">
          <div className="flex justify-between items-end mb-2">
            <h2 className="text-lg font-bold text-slate-800">Your Progress</h2>
            <span className="text-emerald-600 font-bold text-sm">{stats.completed}/{stats.total} Completed</span>
          </div>
          <div className="h-3 w-full bg-slate-200 rounded-full overflow-hidden">
            <div 
              className="h-full bg-gradient-to-r from-emerald-400 to-emerald-600 rounded-full transition-all duration-700 ease-out"
              style={{ width: `${stats.progress}%` }}
            />
          </div>
        </div>

        {/* --- Habits List --- */}
        <div className="space-y-2">
          {habits.length === 0 ? (
            <div className="text-center py-16 bg-white rounded-3xl border border-dashed border-slate-300">
              <div className="inline-flex items-center justify-center w-16 h-16 rounded-full bg-indigo-50 text-indigo-400 mb-4">
                <Activity size={32} />
              </div>
              <h3 className="text-lg font-bold text-slate-700 mb-1">No habits yet</h3>
              <p className="text-slate-400 max-w-xs mx-auto mb-6">Start building your streak today by adding your first habit.</p>
              <button 
                onClick={() => setIsAddModalOpen(true)}
                className="px-6 py-2 bg-indigo-600 hover:bg-indigo-700 text-white rounded-full font-bold transition-colors shadow-lg shadow-indigo-200"
              >
                Create Habit
              </button>
            </div>
          ) : (
            habits.map(habit => (
              <HabitCard key={habit.id} habit={habit} />
            ))
          )}
        </div>

      </main>

      {/* --- Floating Action Button --- */}
      <button
        onClick={() => setIsAddModalOpen(true)}
        className="fixed bottom-8 right-8 md:bottom-12 md:right-[calc(50%-320px)] w-16 h-16 bg-indigo-600 text-white rounded-full shadow-xl hover:bg-indigo-700 hover:scale-105 active:scale-95 transition-all duration-200 flex items-center justify-center z-50 group"
      >
        <Plus size={32} strokeWidth={2.5} className="group-hover:rotate-90 transition-transform duration-300" />
      </button>

      {/* --- Add Habit Modal --- */}
      {isAddModalOpen && (
        <div className="fixed inset-0 z-50 flex items-end md:items-center justify-center p-4 sm:p-6">
          <div 
            className="absolute inset-0 bg-slate-900/40 backdrop-blur-sm transition-opacity" 
            onClick={() => setIsAddModalOpen(false)}
          />
          <div className="relative w-full max-w-md bg-white rounded-3xl p-6 shadow-2xl transform transition-all animate-in slide-in-from-bottom-10 fade-in duration-300">
            <h2 className="text-2xl font-black text-slate-800 mb-6">New Habit</h2>
            
            <form onSubmit={addHabit}>
              <div className="space-y-4 mb-8">
                <div>
                  <label className="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">Habit Name</label>
                  <input
                    type="text"
                    value={newHabitTitle}
                    onChange={(e) => setNewHabitTitle(e.target.value)}
                    placeholder="e.g., Read for 15 mins"
                    className="w-full px-4 py-3 bg-slate-50 border border-slate-200 rounded-xl focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all font-medium text-slate-800 placeholder:text-slate-400"
                    autoFocus
                  />
                </div>

                <div>
                  <label className="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">Category</label>
                  <div className="grid grid-cols-4 gap-2">
                    {Object.keys(ICONS).slice(0, 8).map(cat => {
                      const Icon = ICONS[cat];
                      const isSelected = newHabitCategory === cat;
                      const activeColor = COLORS[cat];
                      
                      return (
                        <button
                          key={cat}
                          type="button"
                          onClick={() => setNewHabitCategory(cat)}
                          className={`
                            p-3 rounded-xl flex items-center justify-center transition-all duration-200
                            ${isSelected 
                              ? `${activeColor} text-white shadow-md scale-105` 
                              : 'bg-slate-50 text-slate-400 hover:bg-slate-100 hover:text-slate-600'
                            }
                          `}
                          title={cat.charAt(0).toUpperCase() + cat.slice(1)}
                        >
                          <Icon size={20} />
                        </button>
                      );
                    })}
                  </div>
                </div>
              </div>

              <div className="flex gap-3">
                <button
                  type="button"
                  onClick={() => setIsAddModalOpen(false)}
                  className="flex-1 py-3.5 rounded-xl font-bold text-slate-500 hover:bg-slate-50 transition-colors"
                >
                  Cancel
                </button>
                <button
                  type="submit"
                  disabled={!newHabitTitle.trim()}
                  className="flex-1 py-3.5 rounded-xl font-bold bg-indigo-600 text-white shadow-lg shadow-indigo-200 hover:bg-indigo-700 disabled:opacity-50 disabled:cursor-not-allowed transition-all"
                >
                  Create Habit
                </button>
              </div>
            </form>
          </div>
        </div>
      )}

    </div>
  );
}
